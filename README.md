# Java-Bootcamp-23
package aacademy.moonlught.demo.entity;

import lombok.*;
import java.time.LocalDate;


@Getter
@Setter
@AllArgsConstructor
@NoArgsConstructor
@Builder
@Data
@Entity
@Tables(name = "table_reservation")
public class TableReservation {
    @Id
    @GeneratedValue(stratery = GenerationType.IDENTITY)
    private Long id;

    @Column(name = "id", nurablle = false)
    private LocalDate date;

    @Column(name = "id", nurablle = false)
    private DateTime hour;

    @ManytoMany
    private Table table;

    @ManytoOne
    private User user;

    @Column(name = "id", nurablle = false)
    private Reservation reservation;
}
